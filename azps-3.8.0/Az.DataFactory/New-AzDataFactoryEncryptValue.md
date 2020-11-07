---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847232"
---
# <span data-ttu-id="f5898-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="f5898-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="f5898-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5898-102">SYNOPSIS</span></span>
<span data-ttu-id="f5898-103">Verschlüsselt vertrauliche Daten.</span><span class="sxs-lookup"><span data-stu-id="f5898-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="f5898-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5898-104">SYNTAX</span></span>

### <span data-ttu-id="f5898-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5898-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5898-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f5898-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5898-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5898-107">DESCRIPTION</span></span>
<span data-ttu-id="f5898-108">Das Cmdlet **New-AzDataFactoryEncryptValue** verschlüsselt vertrauliche Daten wie ein Kennwort oder eine Microsoft SQL Server-Verbindungszeichenfolge und gibt einen verschlüsselten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f5898-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="f5898-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5898-109">EXAMPLES</span></span>

### <span data-ttu-id="f5898-110">Beispiel 1: Verschlüsseln einer nicht-ODBC-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f5898-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="f5898-111">Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um die angegebene Verbindungszeichenfolge in ein **SecureString** -Objekt zu konvertieren, und speichert dieses Objekt dann in der Variablen $value.</span><span class="sxs-lookup"><span data-stu-id="f5898-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="f5898-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="f5898-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="f5898-113">Zulässige Werte: SQL Server-oder Oracle-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f5898-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="f5898-114">Der zweite Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5898-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f5898-115">Beispiel 2: Verschlüsseln einer nicht-ODBC-Verbindungszeichenfolge, die die Windows-Authentifizierung verwendet</span><span class="sxs-lookup"><span data-stu-id="f5898-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="f5898-116">Der erste Befehl verwendet **ConvertTo-SecureString** , um die angegebene Verbindungszeichenfolge in ein sicheres Zeichenfolgenobjekt zu konvertieren, und speichert dieses Objekt dann in der $Value Variablen.</span><span class="sxs-lookup"><span data-stu-id="f5898-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="f5898-117">Der zweite Befehl verwendet das Get-Credential-Cmdlet, um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen, und speichert dann das **PSCredential** -Objekt in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f5898-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="f5898-118">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f5898-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="f5898-119">Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5898-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f5898-120">Beispiel 3: Verschlüsseln des Server namens und der Anmeldeinformationen für den Dateisystem-verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="f5898-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="f5898-121">Der erste Befehl verwendet **ConvertTo-SecureString** , um die angegebene Zeichenfolge in eine sichere Zeichenfolge zu konvertieren, und speichert dieses Objekt dann in der $Value Variablen.</span><span class="sxs-lookup"><span data-stu-id="f5898-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="f5898-122">Der zweite Befehl verwendet **Get-Credential** , um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen, und speichert dann das **PSCredential** -Objekt in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f5898-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="f5898-123">Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5898-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f5898-124">Beispiel 4: Verschlüsseln von Anmeldeinformationen für HDFS-verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="f5898-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="f5898-125">Der Befehl **ConvertTo-SecureString** wandelt die angegebene Zeichenfolge in eine sichere Zeichenfolge um.</span><span class="sxs-lookup"><span data-stu-id="f5898-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="f5898-126">Mit dem Befehl " **New-Object** " wird ein PSCredential-Objekt mithilfe der Zeichenfolgen für sicheres Benutzernamen und Kennwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5898-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="f5898-127">Stattdessen können Sie den Befehl **Get-Credential** verwenden, um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen und dann das zurückgegebene **PSCredential** -Objekt in der $Credential-Variable zu speichern, wie in den vorherigen Beispielen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5898-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="f5898-128">Der Befehl **New-AzDataFactoryEncryptValue** erstellt einen verschlüsselten Wert für das Objekt, das in $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5898-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f5898-129">Beispiel 5: Verschlüsseln von Anmeldeinformationen für ODBC-verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="f5898-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="f5898-130">Der Befehl **ConvertTo-SecureString** wandelt die angegebene Zeichenfolge in eine sichere Zeichenfolge um.</span><span class="sxs-lookup"><span data-stu-id="f5898-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="f5898-131">Der Befehl **New-AzDataFactoryEncryptValue** erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5898-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="f5898-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5898-132">PARAMETERS</span></span>

### <span data-ttu-id="f5898-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f5898-133">-AuthenticationType</span></span>
<span data-ttu-id="f5898-134">Gibt den Authentifizierungstyp an, der für die Verbindung mit der Datenquelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5898-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="f5898-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f5898-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f5898-136">Windows</span><span class="sxs-lookup"><span data-stu-id="f5898-136">Windows</span></span>
- <span data-ttu-id="f5898-137">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="f5898-137">Basic</span></span>
- <span data-ttu-id="f5898-138">Anonyme.</span><span class="sxs-lookup"><span data-stu-id="f5898-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-139">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f5898-139">-Credential</span></span>
<span data-ttu-id="f5898-140">Gibt die Windows-Authentifizierungsanmeldeinformationen (Benutzername und Kennwort) an, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f5898-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="f5898-141">Mit diesem Cmdlet werden die hier angegebenen Anmeldeinformationsdaten verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="f5898-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-142">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f5898-142">-Database</span></span>
<span data-ttu-id="f5898-143">Gibt den Datenbanknamen des verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="f5898-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5898-144">-DataFactory</span></span>
<span data-ttu-id="f5898-145">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f5898-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f5898-146">Dieses Cmdlet verschlüsselt Daten für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f5898-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-147">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f5898-147">-DataFactoryName</span></span>
<span data-ttu-id="f5898-148">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="f5898-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5898-149">Dieses Cmdlet verschlüsselt Daten für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f5898-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5898-150">-DefaultProfile</span></span>
<span data-ttu-id="f5898-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f5898-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5898-152">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="f5898-152">-GatewayName</span></span>
<span data-ttu-id="f5898-153">Gibt den Namen des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="f5898-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="f5898-154">Dieses Cmdlet verschlüsselt Daten für das Gateway, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f5898-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-155">-Nicht credentialvalue</span><span class="sxs-lookup"><span data-stu-id="f5898-155">-NonCredentialValue</span></span>
<span data-ttu-id="f5898-156">Gibt den Teil der nicht-Anmeldeinformationen der ODBC-Verbindungszeichenfolge (Open Database Connectivity) an.</span><span class="sxs-lookup"><span data-stu-id="f5898-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="f5898-157">Dieser Parameter ist nur für den ODBC-verknüpften Dienst anwendbar.</span><span class="sxs-lookup"><span data-stu-id="f5898-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5898-158">-ResourceGroupName</span></span>
<span data-ttu-id="f5898-159">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f5898-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5898-160">Dieses Cmdlet verschlüsselt Daten für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f5898-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-161">-Server</span><span class="sxs-lookup"><span data-stu-id="f5898-161">-Server</span></span>
<span data-ttu-id="f5898-162">Gibt den Servernamen des verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="f5898-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-163">-Typ</span><span class="sxs-lookup"><span data-stu-id="f5898-163">-Type</span></span>
<span data-ttu-id="f5898-164">Gibt den verknüpften Diensttyp an.</span><span class="sxs-lookup"><span data-stu-id="f5898-164">Specifies the linked service type.</span></span>
<span data-ttu-id="f5898-165">Mit diesem Cmdlet werden Daten für den Typ des verknüpften Diensts verschlüsselt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f5898-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="f5898-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f5898-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f5898-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="f5898-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="f5898-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="f5898-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="f5898-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="f5898-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="f5898-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="f5898-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="f5898-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5898-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-176">-Wert</span><span class="sxs-lookup"><span data-stu-id="f5898-176">-Value</span></span>
<span data-ttu-id="f5898-177">Gibt den zu verschlüsselenden Wert an.</span><span class="sxs-lookup"><span data-stu-id="f5898-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="f5898-178">Verwenden Sie für einen lokalen SQL Server-verknüpften Dienst und einen lokalen Oracle-verknüpften Dienst eine Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f5898-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="f5898-179">Verwenden Sie für einen lokalen ODBC-verknüpften Dienst den Anmelde Informationsteil der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f5898-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="f5898-180">Verwenden Sie für den verknüpften Dienst im lokalen Dateisystem, wenn das Dateisystem lokal auf dem Gatewaycomputer vorhanden ist, local oder localhost, und wenn sich das Dateisystem auf einem anderen Server als dem Gatewaycomputer befindet, verwenden Sie \\ \\ Servername.</span><span class="sxs-lookup"><span data-stu-id="f5898-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5898-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5898-181">CommonParameters</span></span>
<span data-ttu-id="f5898-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5898-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5898-183">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5898-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5898-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5898-184">INPUTS</span></span>

### <span data-ttu-id="f5898-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f5898-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f5898-186">System. String</span><span class="sxs-lookup"><span data-stu-id="f5898-186">System.String</span></span>

## <span data-ttu-id="f5898-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5898-187">OUTPUTS</span></span>

### <span data-ttu-id="f5898-188">System. String</span><span class="sxs-lookup"><span data-stu-id="f5898-188">System.String</span></span>

## <span data-ttu-id="f5898-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5898-189">NOTES</span></span>
* <span data-ttu-id="f5898-190">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="f5898-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5898-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5898-191">RELATED LINKS</span></span>

[<span data-ttu-id="f5898-192">Neu – AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="f5898-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


