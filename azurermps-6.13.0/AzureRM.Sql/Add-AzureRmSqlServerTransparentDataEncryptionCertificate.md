---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499393"
---
# <span data-ttu-id="c7b63-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c7b63-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="c7b63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7b63-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b63-103">Hinzufügen eines transparenten Daten Verschlüsselungszertifikats für die angegebene SQL Server-Instanz</span><span class="sxs-lookup"><span data-stu-id="c7b63-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7b63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7b63-104">SYNTAX</span></span>

### <span data-ttu-id="c7b63-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7b63-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b63-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7b63-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b63-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7b63-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7b63-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7b63-108">DESCRIPTION</span></span>
<span data-ttu-id="c7b63-109">Das Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate fügt ein transparentes Daten Verschlüsselungszertifikat für die angegebene SQL Server-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7b63-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="c7b63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7b63-110">EXAMPLES</span></span>

### <span data-ttu-id="c7b63-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7b63-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="c7b63-112">Hinzufügen eines DSA-Zertifikats zu einem SQL Server mit dem Namen der Ressourcengruppe und dem SQL Server-Namen</span><span class="sxs-lookup"><span data-stu-id="c7b63-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="c7b63-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c7b63-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="c7b63-114">Hinzufügen eines DSA-Zertifikats zu den Servern mithilfe der Server-Resourcen-unter Verwendung</span><span class="sxs-lookup"><span data-stu-id="c7b63-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="c7b63-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c7b63-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="c7b63-116">Hinzufügen eines DSA-Zertifikats zu allen SQL-Servern in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c7b63-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="c7b63-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7b63-117">PARAMETERS</span></span>

### <span data-ttu-id="c7b63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b63-118">-DefaultProfile</span></span>
<span data-ttu-id="c7b63-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7b63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b63-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7b63-120">-PassThru</span></span>
<span data-ttu-id="c7b63-121">Bei erfolgreicher Ausführung gibt Certificate-Objekt zurück, das hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c7b63-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="c7b63-122">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="c7b63-122">-Password</span></span>
<span data-ttu-id="c7b63-123">Das Kennwort für das transparente Daten Verschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="c7b63-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="c7b63-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="c7b63-124">-PrivateBlob</span></span>
<span data-ttu-id="c7b63-125">Das private BLOB für das transparente Daten Verschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="c7b63-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="c7b63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b63-126">-ResourceGroupName</span></span>
<span data-ttu-id="c7b63-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c7b63-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="c7b63-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="c7b63-128">-ServerName</span></span>
<span data-ttu-id="c7b63-129">Der Server Name</span><span class="sxs-lookup"><span data-stu-id="c7b63-129">The Server Name</span></span>

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

### <span data-ttu-id="c7b63-130">-SQLServer</span><span class="sxs-lookup"><span data-stu-id="c7b63-130">-SqlServer</span></span>
<span data-ttu-id="c7b63-131">Das SQL Server-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="c7b63-131">The sql server input object</span></span>

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

### <span data-ttu-id="c7b63-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b63-132">-SqlServerResourceId</span></span>
<span data-ttu-id="c7b63-133">Die SQL Server-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c7b63-133">The sql server resource id</span></span>

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

### <span data-ttu-id="c7b63-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7b63-134">-Confirm</span></span>
<span data-ttu-id="c7b63-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7b63-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7b63-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7b63-136">-WhatIf</span></span>
<span data-ttu-id="c7b63-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7b63-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7b63-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7b63-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7b63-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b63-139">CommonParameters</span></span>
<span data-ttu-id="c7b63-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b63-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b63-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b63-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b63-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7b63-142">INPUTS</span></span>

### <span data-ttu-id="c7b63-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c7b63-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="c7b63-144">Parameter: SQLServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7b63-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="c7b63-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c7b63-145">System.String</span></span>

## <span data-ttu-id="c7b63-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7b63-146">OUTPUTS</span></span>

### <span data-ttu-id="c7b63-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7b63-147">System.Boolean</span></span>

## <span data-ttu-id="c7b63-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7b63-148">NOTES</span></span>

## <span data-ttu-id="c7b63-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7b63-149">RELATED LINKS</span></span>
