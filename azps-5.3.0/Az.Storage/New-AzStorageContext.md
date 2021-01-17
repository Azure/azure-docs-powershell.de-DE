---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374056"
---
# <span data-ttu-id="a9314-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9314-101">New-AzStorageContext</span></span>

## <span data-ttu-id="a9314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9314-102">SYNOPSIS</span></span>
<span data-ttu-id="a9314-103">Erstellt einen Azure Storage-Kontext.</span><span class="sxs-lookup"><span data-stu-id="a9314-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="a9314-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9314-104">SYNTAX</span></span>

### <span data-ttu-id="a9314-105">OAuthAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9314-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a9314-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="a9314-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a9314-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="a9314-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="a9314-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="a9314-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9314-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="a9314-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a9314-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="a9314-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a9314-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a9314-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a9314-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="a9314-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="a9314-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9314-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="a9314-114">Local Durch</span><span class="sxs-lookup"><span data-stu-id="a9314-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="a9314-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9314-115">DESCRIPTION</span></span>
<span data-ttu-id="a9314-116">Das **Cmdlet "New-AzStorageContext"** erstellt einen Azure Storage-Kontext.</span><span class="sxs-lookup"><span data-stu-id="a9314-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="a9314-117">Die Standardauthentifizierung eines Speicherkontexts ist OAuth (Azure AD), wenn nur der Name des Speicherkontos eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9314-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="a9314-118">Details zur Authentifizierung des Speicherdiensts finden Sie https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services in.</span><span class="sxs-lookup"><span data-stu-id="a9314-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="a9314-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9314-119">EXAMPLES</span></span>

### <span data-ttu-id="a9314-120">Beispiel 1: Erstellen eines Kontexts durch Angeben des Namens und Schlüssels eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a9314-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="a9314-121">Mit diesem Befehl wird ein Kontext für das Konto "ContosoGeneral" erstellt, das den angegebenen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9314-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a9314-122">Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a9314-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="a9314-123">Mit diesem Befehl wird ein Kontext erstellt, der auf der angegebenen Verbindungszeichenfolge für das Konto "ContosoGeneral" basiert.</span><span class="sxs-lookup"><span data-stu-id="a9314-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="a9314-124">Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="a9314-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="a9314-125">Mit diesem Befehl wird ein Kontext für die anonyme Verwendung für das Konto "ContosoGeneral" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9314-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="a9314-126">Der Befehl gibt HTTP als Verbindungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="a9314-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="a9314-127">Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen Entwicklungsspeicherkontos</span><span class="sxs-lookup"><span data-stu-id="a9314-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="a9314-128">Dieser Befehl erstellt einen Kontext mithilfe des lokalen Entwicklungsspeicherkontos.</span><span class="sxs-lookup"><span data-stu-id="a9314-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="a9314-129">Der Befehl gibt den Parameter *"Local"* an.</span><span class="sxs-lookup"><span data-stu-id="a9314-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="a9314-130">Beispiel 5: Container für das lokale Entwicklerspeicherkonto erhalten</span><span class="sxs-lookup"><span data-stu-id="a9314-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="a9314-131">Dieser Befehl erstellt mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das **Get-AzStorageContainer-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="a9314-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a9314-132">Der Befehl ruft den Azure Storage-Container für das lokale Entwicklerspeicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="a9314-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="a9314-133">Beispiel 6: Mehrere Container erhalten</span><span class="sxs-lookup"><span data-stu-id="a9314-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="a9314-134">Der erste Befehl erstellt mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext und speichert diesen Kontext dann in der $Context 01-Variable.</span><span class="sxs-lookup"><span data-stu-id="a9314-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="a9314-135">Der zweite Befehl erstellt einen Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet, und speichert diesen Kontext dann in der $Context 02-Variable.</span><span class="sxs-lookup"><span data-stu-id="a9314-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="a9314-136">Der letzte Befehl ruft die Container für die in $Context 01 und $Context 02 gespeicherten Kontexte mit **"Get-AzStorageContainer" ab.**</span><span class="sxs-lookup"><span data-stu-id="a9314-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="a9314-137">Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="a9314-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="a9314-138">Mit diesem Befehl wird ein Azure Storage-Kontext erstellt, der den angegebenen Speicherendpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="a9314-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="a9314-139">Der Befehl erstellt den Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9314-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a9314-140">Beispiel 8: Erstellen eines Kontexts mit einer bestimmten Umgebung</span><span class="sxs-lookup"><span data-stu-id="a9314-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="a9314-141">Mit diesem Befehl wird ein Azure-Speicherkontext erstellt, der über die angegebene Azure-Umgebung verfügt.</span><span class="sxs-lookup"><span data-stu-id="a9314-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="a9314-142">Der Befehl erstellt den Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9314-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a9314-143">Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="a9314-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="a9314-144">Der erste Befehl generiert ein SAS-Token mithilfe des **Cmdlets "New-AzStorageContainerSASToken"** für den Container "ContosoMain" und speichert dieses Token dann in der $SasToken-Variable.</span><span class="sxs-lookup"><span data-stu-id="a9314-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="a9314-145">Dieses Token ist für Berechtigungen zum Lesen, Hinzufügen, Aktualisieren und Löschen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9314-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="a9314-146">Der zweite Befehl erstellt einen Kontext für das Konto "ContosoGeneral", das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="a9314-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="a9314-147">Der letzte Befehl listet alle blobs auf, die dem Container "ContosoMain" zugeordnet sind, indem der in der Datei gespeicherte Kontext $Context.</span><span class="sxs-lookup"><span data-stu-id="a9314-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="a9314-148">Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth Authentication</span><span class="sxs-lookup"><span data-stu-id="a9314-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="a9314-149">Mit diesem Befehl wird mithilfe der OAuth (Azure AD)-Authentifizierung ein Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9314-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="a9314-150">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9314-150">PARAMETERS</span></span>

### <span data-ttu-id="a9314-151">-Anonym</span><span class="sxs-lookup"><span data-stu-id="a9314-151">-Anonymous</span></span>
<span data-ttu-id="a9314-152">Gibt an, dass mit diesem Cmdlet ein Azure Storage-Kontext für die anonyme Anmeldung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a9314-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9314-153">-ConnectionString</span></span>
<span data-ttu-id="a9314-154">Gibt eine Verbindungszeichenfolge für den Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="a9314-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="a9314-155">-Endpoint</span></span>
<span data-ttu-id="a9314-156">Gibt den Endpunkt für den Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="a9314-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-157">-Environment</span><span class="sxs-lookup"><span data-stu-id="a9314-157">-Environment</span></span>
<span data-ttu-id="a9314-158">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="a9314-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="a9314-159">Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="a9314-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="a9314-160">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-AzEnvironment` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="a9314-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-161">-Local</span><span class="sxs-lookup"><span data-stu-id="a9314-161">-Local</span></span>
<span data-ttu-id="a9314-162">Gibt an, dass dieses Cmdlet mit dem lokalen Entwicklungsspeicherkonto einen Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9314-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a9314-163">-Protocol</span></span>
<span data-ttu-id="a9314-164">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="a9314-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a9314-165">-SasToken</span></span>
<span data-ttu-id="a9314-166">Gibt ein Sasstoken (Shared Access Signature) für den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="a9314-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a9314-167">-StorageAccountKey</span></span>
<span data-ttu-id="a9314-168">Gibt einen Azure Storage-Kontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="a9314-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="a9314-169">Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a9314-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a9314-170">-StorageAccountName</span></span>
<span data-ttu-id="a9314-171">Gibt den Namen eines Azure Storage-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a9314-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="a9314-172">Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a9314-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="a9314-173">-UseConnectedAccount</span></span>
<span data-ttu-id="a9314-174">Gibt an, dass dieses Cmdlet einen Azure -Speicherkontext mit OAuth (Azure AD)-Authentifizierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9314-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="a9314-175">Das Cmdlet verwendet standardmäßig die OAuth-Authentifizierung, wenn keine andere Authentifizierung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a9314-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9314-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9314-176">CommonParameters</span></span>
<span data-ttu-id="a9314-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9314-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9314-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9314-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9314-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9314-179">INPUTS</span></span>

### <span data-ttu-id="a9314-180">System.String</span><span class="sxs-lookup"><span data-stu-id="a9314-180">System.String</span></span>

## <span data-ttu-id="a9314-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9314-181">OUTPUTS</span></span>

### <span data-ttu-id="a9314-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9314-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="a9314-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9314-183">NOTES</span></span>

## <span data-ttu-id="a9314-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9314-184">RELATED LINKS</span></span>

[<span data-ttu-id="a9314-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a9314-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a9314-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a9314-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


