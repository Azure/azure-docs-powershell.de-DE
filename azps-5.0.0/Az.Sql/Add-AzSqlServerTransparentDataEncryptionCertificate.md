---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175410"
---
# <span data-ttu-id="a7135-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a7135-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="a7135-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7135-102">SYNOPSIS</span></span>
<span data-ttu-id="a7135-103">Hinzufügen eines transparenten Daten Verschlüsselungszertifikats für die angegebene SQL Server-Instanz</span><span class="sxs-lookup"><span data-stu-id="a7135-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="a7135-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7135-104">SYNTAX</span></span>

### <span data-ttu-id="a7135-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7135-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7135-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7135-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7135-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7135-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7135-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7135-108">DESCRIPTION</span></span>
<span data-ttu-id="a7135-109">Das Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate fügt ein transparentes Daten Verschlüsselungszertifikat für die angegebene SQL Server-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7135-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="a7135-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7135-110">EXAMPLES</span></span>

### <span data-ttu-id="a7135-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7135-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="a7135-112">Hinzufügen eines DSA-Zertifikats zu einem SQL Server mit dem Namen der Ressourcengruppe und dem SQL Server-Namen</span><span class="sxs-lookup"><span data-stu-id="a7135-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="a7135-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a7135-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="a7135-114">Hinzufügen eines DSA-Zertifikats zu den Servern mithilfe der Server-Resourcen-unter Verwendung</span><span class="sxs-lookup"><span data-stu-id="a7135-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="a7135-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a7135-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="a7135-116">Hinzufügen eines DSA-Zertifikats zu allen SQL-Servern in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a7135-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="a7135-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7135-117">PARAMETERS</span></span>

### <span data-ttu-id="a7135-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7135-118">-DefaultProfile</span></span>
<span data-ttu-id="a7135-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7135-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7135-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7135-120">-PassThru</span></span>
<span data-ttu-id="a7135-121">Bei erfolgreicher Ausführung gibt Certificate-Objekt zurück, das hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7135-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="a7135-122">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="a7135-122">-Password</span></span>
<span data-ttu-id="a7135-123">Das Kennwort für das transparente Daten Verschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="a7135-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="a7135-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="a7135-124">-PrivateBlob</span></span>
<span data-ttu-id="a7135-125">Das private BLOB für das transparente Daten Verschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="a7135-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="a7135-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7135-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7135-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a7135-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="a7135-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="a7135-128">-ServerName</span></span>
<span data-ttu-id="a7135-129">Der Server Name</span><span class="sxs-lookup"><span data-stu-id="a7135-129">The Server Name</span></span>

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

### <span data-ttu-id="a7135-130">-SQLServer</span><span class="sxs-lookup"><span data-stu-id="a7135-130">-SqlServer</span></span>
<span data-ttu-id="a7135-131">Das SQL Server-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="a7135-131">The sql server input object</span></span>

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

### <span data-ttu-id="a7135-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="a7135-132">-SqlServerResourceId</span></span>
<span data-ttu-id="a7135-133">Die SQL Server-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a7135-133">The sql server resource id</span></span>

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

### <span data-ttu-id="a7135-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7135-134">-Confirm</span></span>
<span data-ttu-id="a7135-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7135-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7135-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7135-136">-WhatIf</span></span>
<span data-ttu-id="a7135-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7135-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7135-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7135-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7135-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7135-139">CommonParameters</span></span>
<span data-ttu-id="a7135-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7135-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7135-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7135-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7135-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7135-142">INPUTS</span></span>

### <span data-ttu-id="a7135-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a7135-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="a7135-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a7135-144">System.String</span></span>

## <span data-ttu-id="a7135-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7135-145">OUTPUTS</span></span>

### <span data-ttu-id="a7135-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7135-146">System.Boolean</span></span>

## <span data-ttu-id="a7135-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7135-147">NOTES</span></span>

## <span data-ttu-id="a7135-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7135-148">RELATED LINKS</span></span>
