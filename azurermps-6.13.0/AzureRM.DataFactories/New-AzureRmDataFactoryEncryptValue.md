---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 5de4c34281b2122880a683f070e771dc15d93c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502997"
---
# <span data-ttu-id="9eea9-101">New-AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="9eea9-101">New-AzureRmDataFactoryEncryptValue</span></span>

## <span data-ttu-id="9eea9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9eea9-102">SYNOPSIS</span></span>
<span data-ttu-id="9eea9-103">Verschlüsselt vertrauliche Daten.</span><span class="sxs-lookup"><span data-stu-id="9eea9-103">Encrypts sensitive data.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eea9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eea9-104">SYNTAX</span></span>

### <span data-ttu-id="9eea9-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9eea9-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eea9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9eea9-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eea9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9eea9-107">DESCRIPTION</span></span>
<span data-ttu-id="9eea9-108">Das Cmdlet **New-AzureRmDataFactoryEncryptValue** verschlüsselt vertrauliche Daten wie ein Kennwort oder eine Microsoft SQL Server-Verbindungszeichenfolge und gibt einen verschlüsselten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9eea9-108">The **New-AzureRmDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="9eea9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9eea9-109">EXAMPLES</span></span>

### <span data-ttu-id="9eea9-110">Beispiel 1: Verschlüsseln einer nicht-ODBC-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9eea9-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="9eea9-111">Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um die angegebene Verbindungszeichenfolge in ein **SecureString** -Objekt zu konvertieren, und speichert dieses Objekt dann in der Variablen $value.</span><span class="sxs-lookup"><span data-stu-id="9eea9-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="9eea9-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9eea9-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="9eea9-113">Zulässige Werte: SQL Server-oder Oracle-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9eea9-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="9eea9-114">Der zweite Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9eea9-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="9eea9-115">Beispiel 2: Verschlüsseln einer nicht-ODBC-Verbindungszeichenfolge, die die Windows-Authentifizierung verwendet</span><span class="sxs-lookup"><span data-stu-id="9eea9-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="9eea9-116">Der erste Befehl verwendet **ConvertTo-SecureString** , um die angegebene Verbindungszeichenfolge in ein sicheres Zeichenfolgenobjekt zu konvertieren, und speichert dieses Objekt dann in der $Value Variablen.</span><span class="sxs-lookup"><span data-stu-id="9eea9-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="9eea9-117">Der zweite Befehl verwendet das Get-Credential-Cmdlet, um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen, und speichert dann das **PSCredential** -Objekt in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9eea9-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="9eea9-118">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9eea9-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="9eea9-119">Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9eea9-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="9eea9-120">Beispiel 3: Verschlüsseln des Server namens und der Anmeldeinformationen für den Dateisystem-verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="9eea9-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="9eea9-121">Der erste Befehl verwendet **ConvertTo-SecureString** , um die angegebene Zeichenfolge in eine sichere Zeichenfolge zu konvertieren, und speichert dieses Objekt dann in der $Value Variablen.</span><span class="sxs-lookup"><span data-stu-id="9eea9-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="9eea9-122">Der zweite Befehl verwendet **Get-Credential** , um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen, und speichert dann das **PSCredential** -Objekt in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9eea9-122">The second command uses **Get-Credential** to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="9eea9-123">Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9eea9-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="9eea9-124">Beispiel 4: Verschlüsseln von Anmeldeinformationen für HDFS-verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="9eea9-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="9eea9-125">Der Befehl **ConvertTo-SecureString** wandelt die angegebene Zeichenfolge in eine sichere Zeichenfolge um.</span><span class="sxs-lookup"><span data-stu-id="9eea9-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="9eea9-126">Mit dem Befehl " **New-Object** " wird ein PSCredential-Objekt mithilfe der Zeichenfolgen für sicheres Benutzernamen und Kennwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="9eea9-127">Stattdessen können Sie den Befehl **Get-Credential** verwenden, um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen und dann das zurückgegebene **PSCredential** -Objekt in der $Credential-Variable zu speichern, wie in den vorherigen Beispielen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-127">Instead, you could use the **Get-Credential** command to collect windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="9eea9-128">Der Befehl **New-AzureRmDataFactoryEncryptValue** erstellt einen verschlüsselten Wert für das Objekt, das in $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9eea9-128">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="9eea9-129">Beispiel 5: Verschlüsseln von Anmeldeinformationen für ODBC-verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="9eea9-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="9eea9-130">Der Befehl **ConvertTo-SecureString** wandelt die angegebene Zeichenfolge in eine sichere Zeichenfolge um.</span><span class="sxs-lookup"><span data-stu-id="9eea9-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="9eea9-131">Der Befehl **New-AzureRmDataFactoryEncryptValue** erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9eea9-131">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="9eea9-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eea9-132">PARAMETERS</span></span>

### <span data-ttu-id="9eea9-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="9eea9-133">-AuthenticationType</span></span>
<span data-ttu-id="9eea9-134">Gibt den Authentifizierungstyp an, der für die Verbindung mit der Datenquelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9eea9-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="9eea9-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9eea9-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9eea9-136">Windows</span><span class="sxs-lookup"><span data-stu-id="9eea9-136">Windows</span></span>
- <span data-ttu-id="9eea9-137">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="9eea9-137">Basic</span></span>
- <span data-ttu-id="9eea9-138">Anonyme.</span><span class="sxs-lookup"><span data-stu-id="9eea9-138">Anonymous.</span></span>

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

### <span data-ttu-id="9eea9-139">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eea9-139">-Credential</span></span>
<span data-ttu-id="9eea9-140">Gibt die Windows-Authentifizierungsanmeldeinformationen (Benutzername und Kennwort) an, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9eea9-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="9eea9-141">Mit diesem Cmdlet werden die hier angegebenen Anmeldeinformationsdaten verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-141">This cmdlet encrypts the credential data you specify here.</span></span>

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

### <span data-ttu-id="9eea9-142">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="9eea9-142">-Database</span></span>
<span data-ttu-id="9eea9-143">Gibt den Datenbanknamen des verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-143">Specifies the database name of the linked service.</span></span>

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

### <span data-ttu-id="9eea9-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9eea9-144">-DataFactory</span></span>
<span data-ttu-id="9eea9-145">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9eea9-146">Dieses Cmdlet verschlüsselt Daten für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9eea9-147">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9eea9-147">-DataFactoryName</span></span>
<span data-ttu-id="9eea9-148">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9eea9-149">Dieses Cmdlet verschlüsselt Daten für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9eea9-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eea9-150">-DefaultProfile</span></span>
<span data-ttu-id="9eea9-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9eea9-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eea9-152">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="9eea9-152">-GatewayName</span></span>
<span data-ttu-id="9eea9-153">Gibt den Namen des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="9eea9-154">Dieses Cmdlet verschlüsselt Daten für das Gateway, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eea9-155">-Nicht credentialvalue</span><span class="sxs-lookup"><span data-stu-id="9eea9-155">-NonCredentialValue</span></span>
<span data-ttu-id="9eea9-156">Gibt den Teil der nicht-Anmeldeinformationen der ODBC-Verbindungszeichenfolge (Open Database Connectivity) an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="9eea9-157">Dieser Parameter ist nur für den ODBC-verknüpften Dienst anwendbar.</span><span class="sxs-lookup"><span data-stu-id="9eea9-157">This parameter is applicable only for the ODBC linked service.</span></span>

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

### <span data-ttu-id="9eea9-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eea9-158">-ResourceGroupName</span></span>
<span data-ttu-id="9eea9-159">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9eea9-160">Dieses Cmdlet verschlüsselt Daten für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9eea9-161">-Server</span><span class="sxs-lookup"><span data-stu-id="9eea9-161">-Server</span></span>
<span data-ttu-id="9eea9-162">Gibt den Servernamen des verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-162">Specifies the server name of the linked service.</span></span>

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

### <span data-ttu-id="9eea9-163">-Typ</span><span class="sxs-lookup"><span data-stu-id="9eea9-163">-Type</span></span>
<span data-ttu-id="9eea9-164">Gibt den verknüpften Diensttyp an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-164">Specifies the linked service type.</span></span>
<span data-ttu-id="9eea9-165">Mit diesem Cmdlet werden Daten für den Typ des verknüpften Diensts verschlüsselt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9eea9-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="9eea9-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9eea9-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9eea9-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="9eea9-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="9eea9-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="9eea9-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="9eea9-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="9eea9-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="9eea9-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="9eea9-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="9eea9-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eea9-175">OnPremisesSybaseLinkedService</span></span>

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

### <span data-ttu-id="9eea9-176">-Wert</span><span class="sxs-lookup"><span data-stu-id="9eea9-176">-Value</span></span>
<span data-ttu-id="9eea9-177">Gibt den zu verschlüsselenden Wert an.</span><span class="sxs-lookup"><span data-stu-id="9eea9-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="9eea9-178">Verwenden Sie für einen lokalen SQL Server-verknüpften Dienst und einen lokalen Oracle-verknüpften Dienst eine Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9eea9-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="9eea9-179">Verwenden Sie für einen lokalen ODBC-verknüpften Dienst den Anmelde Informationsteil der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9eea9-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="9eea9-180">Verwenden Sie für den verknüpften Dienst im lokalen Dateisystem, wenn das Dateisystem lokal auf dem Gatewaycomputer vorhanden ist, local oder localhost, und wenn sich das Dateisystem auf einem anderen Server als dem Gatewaycomputer befindet, verwenden Sie \\ \\ Servername.</span><span class="sxs-lookup"><span data-stu-id="9eea9-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

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

### <span data-ttu-id="9eea9-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eea9-181">CommonParameters</span></span>
<span data-ttu-id="9eea9-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eea9-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eea9-183">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eea9-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eea9-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9eea9-184">INPUTS</span></span>

### <span data-ttu-id="9eea9-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9eea9-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9eea9-186">System. String</span><span class="sxs-lookup"><span data-stu-id="9eea9-186">System.String</span></span>

## <span data-ttu-id="9eea9-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9eea9-187">OUTPUTS</span></span>

### <span data-ttu-id="9eea9-188">System. String</span><span class="sxs-lookup"><span data-stu-id="9eea9-188">System.String</span></span>

## <span data-ttu-id="9eea9-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="9eea9-189">NOTES</span></span>
* <span data-ttu-id="9eea9-190">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="9eea9-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9eea9-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9eea9-191">RELATED LINKS</span></span>

[<span data-ttu-id="9eea9-192">Neu – AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="9eea9-192">New-AzureRmDataFactoryEncryptValue</span></span>](./New-AzureRmDataFactoryEncryptValue.md)


