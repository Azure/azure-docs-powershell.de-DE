---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296224"
---
# <span data-ttu-id="d94b7-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d94b7-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="d94b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d94b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d94b7-103">Fügt ein transparentes Datenverschlüsselungszertifikat für die angegebene SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="d94b7-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="d94b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d94b7-104">SYNTAX</span></span>

### <span data-ttu-id="d94b7-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d94b7-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94b7-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d94b7-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94b7-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d94b7-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94b7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d94b7-108">DESCRIPTION</span></span>
<span data-ttu-id="d94b7-109">Die Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate fügt ein transparentes Datenverschlüsselungszertifikat für die angegebene SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="d94b7-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="d94b7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d94b7-110">EXAMPLES</span></span>

### <span data-ttu-id="d94b7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d94b7-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="d94b7-112">Hinzufügen eines TDE-Zertifikats zu einem Sql Server mithilfe des Ressourcengruppennamens und SQL Server Namen</span><span class="sxs-lookup"><span data-stu-id="d94b7-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="d94b7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d94b7-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="d94b7-114">Hinzufügen eines TDE-Zertifikats zu den Servern mit server resourceId</span><span class="sxs-lookup"><span data-stu-id="d94b7-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="d94b7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d94b7-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="d94b7-116">Hinzufügen eines TDE-Zertifikats zu allen SQL-Servern in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d94b7-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="d94b7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d94b7-117">PARAMETERS</span></span>

### <span data-ttu-id="d94b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94b7-118">-DefaultProfile</span></span>
<span data-ttu-id="d94b7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d94b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d94b7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d94b7-120">-PassThru</span></span>
<span data-ttu-id="d94b7-121">Gibt bei erfolgreicher Ausführung das hinzugefügte Zertifikatobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d94b7-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="d94b7-122">-Password</span><span class="sxs-lookup"><span data-stu-id="d94b7-122">-Password</span></span>
<span data-ttu-id="d94b7-123">Das Kennwort für das Zertifikat zur transparenten Datenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d94b7-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="d94b7-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="d94b7-124">-PrivateBlob</span></span>
<span data-ttu-id="d94b7-125">Das private BLOB für transparente Datenverschlüsselungszertifikate</span><span class="sxs-lookup"><span data-stu-id="d94b7-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="d94b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="d94b7-127">Der Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d94b7-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="d94b7-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d94b7-128">-ServerName</span></span>
<span data-ttu-id="d94b7-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="d94b7-129">The Server Name</span></span>

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

### <span data-ttu-id="d94b7-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="d94b7-130">-SqlServer</span></span>
<span data-ttu-id="d94b7-131">Das Sql Server-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="d94b7-131">The sql server input object</span></span>

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

### <span data-ttu-id="d94b7-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="d94b7-132">-SqlServerResourceId</span></span>
<span data-ttu-id="d94b7-133">Die SQL Server-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d94b7-133">The sql server resource id</span></span>

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

### <span data-ttu-id="d94b7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d94b7-134">-Confirm</span></span>
<span data-ttu-id="d94b7-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d94b7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94b7-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d94b7-136">-WhatIf</span></span>
<span data-ttu-id="d94b7-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d94b7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94b7-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d94b7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94b7-139">CommonParameters</span></span>
<span data-ttu-id="d94b7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94b7-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d94b7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94b7-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d94b7-142">INPUTS</span></span>

### <span data-ttu-id="d94b7-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d94b7-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="d94b7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d94b7-144">System.String</span></span>

## <span data-ttu-id="d94b7-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d94b7-145">OUTPUTS</span></span>

### <span data-ttu-id="d94b7-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d94b7-146">System.Boolean</span></span>

## <span data-ttu-id="d94b7-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d94b7-147">NOTES</span></span>

## <span data-ttu-id="d94b7-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d94b7-148">RELATED LINKS</span></span>
